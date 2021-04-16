---
description: В этом разделе описывается внутренняя структура библиотеки Директксмас.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Внутренние библиотеки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccac708934c393a526fdb46d73f819d6557107f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692619"
---
# <a name="library-internals"></a>Внутренние библиотеки

В этом разделе описывается внутренняя структура библиотеки Директксмас.

-   [Соглашения о вызовах](#calling-conventions)
-   [Эквивалентность типов библиотеки графики](#graphics-library-type-equivalence)
-   [Глобальные константы в библиотеке Директксмас](#global-constants-in-the-directxmath-library)
-   [Windows SSE и SSE2](#windows-sse-versus-sse2)
-   [Варианты подпрограмм](#routine-variants)
-   [Несогласованность платформ](#platform-inconsistencies)
-   [Расширения для конкретной платформы](#platform-specific-extensions)
-   [См. также](#related-topics)

## <a name="calling-conventions"></a>Соглашения о вызовах

Чтобы повысить уровень переносимости и оптимизировать структуру данных, необходимо использовать соответствующие соглашения о вызовах для каждой платформы, поддерживаемой библиотекой Директксмас. В частности, при передаче объектов [**ксмвектор**](xmvector-data-type.md) в качестве параметров, которые определены как выравниваемая по 16-байтовой границе, существуют различные наборы требований к вызову в зависимости от целевой платформы.

**Для 32-разрядной версии Windows**

Для 32-разрядных систем Windows существует два соглашения о вызовах для эффективной передачи значений [ \_ \_ M128](/cpp/cpp/m128) (которые реализуют [**ксмвектор**](xmvector-data-type.md) на этой платформе). Стандартом является [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), который может передавать первые три значения [ \_ \_ M128](/cpp/cpp/m128) (экземпляры **ксмвектор** ) в качестве аргументов в функцию в регистре *SSE/SSE2* . [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx) передает оставшиеся аргументы через стек.

Новые компиляторы Microsoft Visual Studio поддерживают новое соглашение о вызовах, \_ \_ векторкалл, которое может передавать до шести значений [ \_ \_ M128](/cpp/cpp/m128) (экземпляров [**ксмвектор**](xmvector-data-type.md) ) в качестве аргументов функции в регистре *SSE/SSE2* . При наличии достаточного места он также может передавать разнородные статистические выражения (также известные как [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) через регистры *SSE/SSE2* .

**Для 64-разрядных выпусков Windows**

Для 64-разрядных систем Windows доступно два соглашения о вызовах для эффективной передачи значений [ \_ \_ M128](/cpp/cpp/m128) . Стандартом является [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), который передает все значения [ \_ \_ M128](/cpp/cpp/m128) в стеке.

Более новые компиляторы Visual Studio поддерживают \_ \_ соглашение о вызовах векторкалл, которое может передавать до шести значений [ \_ \_ M128](/cpp/cpp/m128) (экземпляров [**ксмвектор**](xmvector-data-type.md) ) в качестве аргументов функции в регистре *SSE/SSE2* . При наличии достаточного места он также может передавать разнородные статистические выражения (также известные как [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) через регистры *SSE/SSE2* .

**Для Windows RT**

Операционная система Windows RT поддерживает передачу первых четырех \_ \_ значений N128 (экземпляров [**ксмвектор**](xmvector-data-type.md) ) в регистре.

**Решение Директксмас**

Псевдонимы **фксмвектор**, **гксмвектор**, **хксмвектор** и **кксмвектор** поддерживают следующие соглашения:

-   Используйте псевдоним **фксмвектор** для передачи первых трех экземпляров [**ксмвектор**](xmvector-data-type.md) , используемых в качестве аргументов функции.
-   Используйте псевдоним **гксмвектор** для передачи 4-го экземпляра [**ксмвектор**](xmvector-data-type.md) , используемого в качестве аргумента функции.
-   Используйте псевдоним **хксмвектор** для передачи 5-и шестого экземпляров [**ксмвектор**](xmvector-data-type.md) , используемого в качестве аргумента функции. Дополнительные сведения о дополнительных вопросах см. в \_ \_ документации по векторкалл.
-   Используйте псевдоним **кксмвектор** для передачи последующих экземпляров [**ксмвектор**](xmvector-data-type.md) , используемых в качестве аргументов.

> [!Note]  
> Для выходных параметров всегда используйте КСМВЕКТОР \* или ксмвектор& и игнорируйте их по отношению к предыдущим правилам для входных параметров.

 

Из-за ограничений \_ \_ векторкалл не рекомендуется использовать **гксмвектор** или **хксмвектор** для конструкторов C++. Просто используйте **фксмвектор** для первых трех значений [**ксмвектор**](xmvector-data-type.md) , а затем используйте **кксмвектор** для остальных.

Псевдонимы **фксмматрикс** и **кксмматрикс** помогают использовать преимущества аргумента Хва, передавая \_ \_ векторкалл.

-   Используйте псевдоним **фксмматрикс** для передачи первого [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) в качестве аргумента функции. Предполагается, что у вас нет более двух аргументов **фксмвектор** или более двух аргументов float, Double или **фксмвектор** для "правого" матрицы. Дополнительные сведения о дополнительных вопросах см. в \_ \_ документации по векторкалл.
-   В противном случае используйте псевдоним **кксмматрикс** .

Из-за ограничений \_ \_ векторкалл рекомендуется никогда не использовать **фксмматрикс** для конструкторов C++. Просто используйте **кксмматрикс**.

Помимо псевдонимов типов необходимо также использовать \_ заметку XM каллконв, чтобы убедиться, что функция использует соответствующее соглашение о вызовах ( \_ \_ fastcall и \_ \_ векторкалл) на основе компилятора и архитектуры. Из-за ограничений \_ \_ векторкалл не рекомендуется использовать XM \_ каллконв для конструкторов C++.

Ниже приведены примеры объявлений, иллюстрирующих это соглашение:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Для поддержки этих соглашений о вызовах эти псевдонимы типов определяются следующим образом (параметры должны передаваться компилятору для их учета при передаче в регистре):

**Для 32-разрядных приложений Windows**

При использовании \_ \_ fastcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



При использовании \_ \_ векторкалл:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Для 64-разрядных собственных приложений Windows**

При использовании \_ \_ fastcall:


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



При использовании \_ \_ векторкалл:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Windows RT**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Хотя все функции объявляются встроенным образом и во многих случаях компилятору не нужно использовать соглашения о вызовах для этих функций, бывают случаи, когда компилятор может решить, что это более эффективно, чем встраивание функции, и в таких случаях нам требуется наилучшее соглашение о вызовах для каждой платформы.

 

## <a name="graphics-library-type-equivalence"></a>Эквивалентность типов библиотеки графики

Для поддержки использования библиотеки Директксмас многие типы и структуры библиотек Директксмас эквивалентны реализациям Windows типов **D3DDECLTYPE** и **D3DFORMAT** , а также типам [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) . 

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | \_Формат DXGI                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | \_Формат DXGI \_ R8G8 \_ Синт                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (только Xbox)                                                        | D3DFMT \_ x8x8x8x8                                              | \_Формат DXGI \_ x8x8x8x8 \_ Синт                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | \_Формат DXGI \_ R8G8 \_ снорм                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (только Xbox)                                                       | D3DFMT \_ x8x8x8x8                                              | \_Формат DXGI \_ x8x8x8x8 \_ снорм                                                                                                                                                                           |
| [**ксмколор**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | \_Формат DXGI \_ B8G8R8A8 \_ UNORM (DXGI 1.1 +)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (только Xbox)                                                         | D3DDECLTYPE \_ DEC3 (только Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (только Xbox)                                                        | D3DDECLTYPE \_ DEC3N (только Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | \_Формат DXGI \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | \_Формат DXGI \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | \_Формат DXGI \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | \_Формат DXGI \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | \_Формат DXGI \_ R11G11B10 \_ float                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | \_Формат DXGI \_ R9G9B9E5 \_ шаредексп                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | \_Формат DXGI \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | \_Формат DXGI \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | \_Формат DXGI \_ R16G16 \_ float                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | \_Формат DXGI \_ R16G16B16A16 \_ float                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | \_Формат DXGI \_ R32G32 \_ Синт                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | \_Формат DXGI \_ R32G32B32 \_ Синт                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | \_Формат DXGI \_ R32G32B32A32 \_ Синт                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | \_Формат DXGI \_ R16G16 \_ Синт                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | \_Формат DXGI \_ R16G16 \_ снорм                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | \_Формат DXGI \_ R16G16B16A16 \_ Синт                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | \_Формат DXGI \_ R16G16B16A16 \_ снорм                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | \_Формат DXGI \_ R8G8 \_ uint                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | \_Формат DXGI \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | \_Формат DXGI \_ R32G32 \_ uint                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | \_Формат DXGI \_ R32G32B32 \_ uint                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | \_Формат DXGI \_ R32G32B32A32 \_ uint                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | \_Формат DXGI \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | \_Формат DXGI \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | \_Формат DXGI \_ x8x8x8x8 \_ uint                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | \_Формат DXGI \_ x8x8x8x8 \_ UNORM<br/> В \_ формате DXGI \_ R10G10B10 \_ XR \_ смещение \_ a2 \_ UNORM (используйте [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) и [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)).<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (только Xbox)<br/> D3DDECLTYPE \_ UDEC3 (только Xbox)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | \_Формат DXGI \_ R10G10B10A2 \_ uint                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (только Xbox)<br/> D3DDECLTYPE \_ UDEC3N (только Xbox)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | \_Формат DXGI \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | \_Формат DXGI \_ B4G4R4A4 \_ UNORM (DXGI 1.2 +)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | \_Формат DXGI \_ R16G16 \_ uint                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | \_Формат DXGI \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (только Xbox)                                                      | D3DFMT \_ x16x16x16x16                                          | \_Формат DXGI \_ R16G16B16A16 \_ uint                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | \_Формат DXGI \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Глобальные константы в библиотеке Директксмас

Чтобы уменьшить размер сегмента данных, Библиотека Директксмас использует макрос [ксмглобалконст](xmglobalconst.md) для использования ряда глобальных внутренних констант в своей реализации. По соглашению такие внутренние глобальные константы имеют префикс **g \_ XM**. Как правило, они являются одним из следующих типов: [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORF32**](xmvectorf32-data-type.md)или **XMVECTORI32**.

Эти внутренние глобальные константы могут быть изменены в будущих редакциях библиотеки Директксмас. Используйте открытые функции, которые инкапсулируют константы, если это возможно, а не непосредственное использование глобальных значений **g \_ XM** . Вы также можете объявить собственные глобальные константы с помощью [ксмглобалконст](xmglobalconst.md).

## <a name="windows-sse-versus-sse2"></a>Windows SSE и SSE2

Набор инструкций SSE обеспечивает поддержку только для векторов с плавающей запятой одиночной точности. Директксмас должен использовать набор инструкций SSE2, чтобы обеспечить поддержку целочисленных векторов. SSE2 поддерживается всеми процессорами Intel, начиная с выпуска Pentium 4, всех процессоров AMD K8 и более поздних версий и всех процессоров с поддержкой x64.

> [!Note]  
> Для Windows 8 для x86 требуется поддержка SSE2. Для всех версий Windows x64 требуется поддержка SSE2. Windows RT (также известная как Windows on ARM) требует ARM \_ Neon.

 

## <a name="routine-variants"></a>Варианты подпрограмм

Существует несколько вариантов функций Директксмас, упрощающих работу:

-   Функции сравнения для создания сложного условного ветвления на основе меньшего количества операций сравнения векторов. Имена этих функций заканчиваются на "R", например XMVector3InBoundsR. Функции возвращают запись сравнения в виде возвращаемого значения UINT или в качестве параметра с параметром UINT out. Для проверки значения можно использовать макросы **ксмкомпарисион \** _.
-   Пакетные функции для выполнения операций в пакетном режиме над большими векторными массивами. Имена этих функций заканчиваются на "Stream", например, [_ *XMVector3TransformStream* *](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream). Функции работают с массивом входов и создают массив выходов. Как правило, они принимают входной и выходной шаг.
-   Функции оценки, которые реализуют более быструю оценку вместо более медленных, более точных результатов. Имена этих функций заканчиваются на "EST", например [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest). Качество и производительность, влияющие на оценку использования оценки, отличаются от платформы к платформе, но мы рекомендуем использовать варианты оценки для кода, чувствительного к производительности.

## <a name="platform-inconsistencies"></a>Несогласованность платформ

Библиотека Директксмас предназначена для использования в графических приложениях и играх с учетом производительности. Таким образом, реализация разработана для оптимальной скорости выполнения обычной обработки на всех поддерживаемых платформах. Результаты на условиях границы, особенно те, которые создают специальные объекты с плавающей запятой, скорее всего, будут отличаться от целевых к целевым. Это поведение также зависит от других параметров времени выполнения, таких как управляющее слово x87 для целевого объекта Windows 32-bit без встроенных функций или управляющего слова SSE для Windows 32-bit и 64-bit. Кроме того, в условиях границ между различными поставщиками ЦП будут обнаружены различия.

Не используйте Директксмас в научных и других приложениях, если точность числовых значений является первостепенное. Кроме того, это ограничение отражается в недостатке поддержки двойного или другого вычисления с высокой точностью.

> [!Note]  
> В \_ XM \_ нет \_ встроенных \_ путей к коду, обычно написанных для обеспечения соответствия, а не производительности. Результаты их границ также будут разными.

 

## <a name="platform-specific-extensions"></a>Расширения для конкретной платформы

Библиотека Директксмас предназначена для упрощения поддержки C++ SIMD-программирования, обеспечивающей отличную поддержку платформ x86, x64 и Windows RT с помощью широко поддерживаемых встроенных инструкций (SSE2 и ARM-NEON).

Однако бывают случаи, когда инструкции, относящиеся к конкретной платформе, могут оказаться полезными. Из-за способа реализации Директксмас во многих случаях довольно просто использовать типы Директксмас непосредственно в стандартных встроенных инструкциях, поддерживаемых компилятором, и использовать Директксмас в качестве резервного пути для платформ, которые не поддерживают расширенную инструкцию.

Например, ниже приведен упрощенный пример использования инструкции по использованию SSE 4,1 Dot-Product. Обратите внимание, что необходимо явно защитить путь кода, чтобы избежать создания исключений недопустимых инструкций во время выполнения. Убедитесь, что пути кода достаточно существенны, чтобы вычислить дополнительную стоимость ветвления, сложность поддержки нескольких путей кода и т. д.


```
#include <windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
   __cpuid( CPUInfo, 0 );

   if ( CPUInfo[0] >= 1 )
   {
       __cpuid(CPUInfo, 1 );
 
       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ... 

   return 0;
}
```



Дополнительные сведения о расширениях для конкретных платформ см. в следующих статьях:

<dl>

[Директксмас: SSE, SSE2 и ARM-NEON](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[Директксмас: SSE3 и SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[Директксмас: SSE 4.1 и SSE 4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[Директксмас: AVX](https://walbourn.github.io/directxmath-avx/)  
[Директксмас: F16C и FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[Директксмас: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[Директксмас: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Директксмас по программированию](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
