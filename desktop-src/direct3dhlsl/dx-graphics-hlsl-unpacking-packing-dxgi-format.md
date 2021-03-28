---
title: Распаковка и упаковка DXGI_FORMAT для изменения изображения In-Place
description: Файл D3DX \_ дксгиформатконверт. inl содержит функции преобразования встроенного формата, которые можно использовать в шейдере вычислений или шейдере пикселей на оборудовании Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329072"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Распаковка и \_ формат упаковки для редактирования образа In-Place

Файл D3DX \_ дксгиформатконверт. inl содержит функции преобразования встроенного формата, которые можно использовать в шейдере вычислений или шейдере пикселей на оборудовании Direct3D 11. Эти функции можно использовать в приложении для одновременного чтения и записи текстуры. Это значит, что можно выполнять редактирование изображений на месте. Чтобы использовать эти функции преобразования встроенного формата, включите в \_ приложение файл D3DX дксгиформатконверт. inl.

Неупорядоченное представление доступа Direct3D 11 (UAV) ресурса Texture1D, Texture2D или Texture3D поддерживает чтение и запись в память из шейдера вычислений или шейдера пикселей. Однако Direct3D 11 поддерживает одновременно чтение из формата R32 uint и запись в него только в формате этой \_ \_ \_ текстуры. Например, Direct3D 11 не поддерживает одновременно чтение из других и запись в другие, более полезные форматы, например, в формате DXGI \_ \_ R8G8B8A8 \_ UNORM. Можно использовать только UAV для записи произвольного доступа в такие форматы, или можно использовать только шейдер представление ресурсов (SRV) для чтения произвольного доступа из таких других форматов. Оборудование для преобразования формата недоступно для одновременного чтения из таких форматов и записи в них.

Тем не менее вы по-прежнему можете одновременно выполнять операции чтения и записи в таких форматах, применяя текстуру к формату R32 uint в формате DXGI \_ \_ \_ , при создании UAV, если исходный формат ресурса поддерживает приведение к \_ формату DXGI \_ R32 \_ uint. В большинстве 32 форматов элементов поддерживается приведение к \_ формату DXGI \_ R32 \_ uint. Путем приведения текстуры к формату \_ R32 uint в формате DXGI \_ \_ , при создании UAV можно одновременно выполнять операции чтения и записи в текстуру, если шейдер выполняет распаковку в ручном формате для чтения и упаковки при записи.

Преимуществом приведения текстуры к формату \_ \_ R32 uint формата DXGI \_ является то, что позже можно будет использовать соответствующий формат (например, в \_ формате DXGI \_ R16G16 \_ float) с другими представлениями на той же текстуре, например представления целевого объекта отрисовки (RTVs) или СРВС. Таким образом, оборудование может выполнять Стандартный автоматический распаковки и упаковки, может выполнять фильтрацию текстур и т. д. в случае отсутствия ограничений на оборудование.

В следующем сценарии требуется, чтобы приложение выполнило следующую последовательность действий для редактирования изображений на месте.

Предположим, вы хотите создать текстуру, на которой можно использовать шейдер пикселей или шейдер для выполнения редактирования на месте, и необходимо, чтобы данные текстуры хранились в формате, который является потомком одного из следующих форматов, не имеющих тип:

-   \_Формат DXGI \_ R10G10B10A2 \_ тип
-   \_Формат DXGI \_ R8G8B8A8 \_ тип
-   \_Формат DXGI \_ B8G8R8A8 \_ тип
-   \_Формат DXGI \_ B8G8R8X8 \_ тип
-   \_Формат DXGI \_ R16G16 \_ тип

Например, формат DXGI \_ \_ R10G10B10A2 UNORM Format \_ является потомком \_ формата DXGI \_ R10G10B10A2 \_ format. Таким образом, \_ Формат DXGI \_ R10G10B10A2 \_ UNORM поддерживает шаблон использования, описанный в следующей последовательности. Форматы, которые \_ \_ относятся к формату R32 \_ без типов, такие как \_ Формат DXGI \_ R32 float, просты в поддержке, \_ не требуя использования справки по преобразованию формата, описанной в следующей последовательности.

**Выполнение редактирования изображений на месте**

1.  Создайте текстуру с соответствующим форматом, зависимым от типа, который указан в предыдущем сценарии, вместе с необходимыми флагами привязки, такими как D3D11 \_ BIND \_ неупорядоченный \_ доступ \| D3D11 \_ BIND \_ \_ Resource Shader.
2.  Для редактирования изображений на месте создайте UAV с \_ \_ \_ форматом DXGI R32 uint. API Direct3D 11 обычно не допускает приведение между различными форматами семейства. Однако API Direct3D 11 создает исключение с форматом DXGI \_ \_ R32 \_ uint Format.
3.  В выстроителе вычислений или шейдере пикселей используйте подходящий пакет встроенного формата и функции распаковки, которые предоставляются в \_ файле D3DX дксгиформатконверт. inl. Например, предположим, что \_ Формат DXGI \_ R32 \_ uint UAV для текстуры действительно содержит формат DXGI \_ \_ R10G10B10A2 \_ UNORM-Format Data. После того как приложение считывает значение uint из UAV в шейдер, оно должно вызвать следующую функцию для распаковки формата текстуры:

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    Затем, чтобы записать данные в UAV в том же шейдере, приложение вызывает следующую функцию для упаковки данных шейдера в uint, которые приложение может записать в UAV:

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  Затем приложение может создать другие представления, например СРВС, с требуемым форматом. Например, приложение может создать SRV с \_ \_ \_ форматом DXGI R10G10B10A2 UNORM, если ресурс был создан как \_ Формат DXGI \_ R10G10B10A2 Type без \_ типа. Когда шейдер получает доступ к этой SRV-записи, оборудование может выполнять автоматическое преобразование типов обычным образом.

> [!Note]  
> Если шейдер должен выполнять запись только в UAV или считывать как SRV, ни одно из этого преобразования не требуется, так как можно использовать полностью типизированный Уавс или СРВС. Функции преобразования формата, предоставляемые в D3DX \_ дксгиформатконверт. inl, потенциально полезны только в том случае, если требуется выполнить одновременное чтение из UAV текстуры и запись в него.

 

Ниже приведен список функций преобразования формата, которые включены в \_ файл D3DX дксгиформатконверт. inl. Эти функции классифицируются по \_ формату DXGI, который они распаковать и упаковать. Каждый из поддерживаемых форматов в порядке убывания из одного из форматов без типа, перечисленных в предыдущем сценарии, и поддерживает приведение к \_ формату DXGI \_ R32 \_ uint в виде UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>\_Формат DXGI \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>\_Формат DXGI \_ R10G10B10A2 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>\_Формат DXGI \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>\_Формат DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> \_Функция неточного типа использует инструкции шейдера, которые не имеют достаточно большой точности для получения точного ответа. Альтернативная функция использует таблицу подстановки, хранящуюся в шейдере, чтобы обеспечить точное преобразование с плавающей запятой SRGB->.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>\_Формат DXGI \_ R8G8B8A8 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>\_Формат DXGI \_ R8G8B8A8 \_ снорм
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Формат DXGI \_ R8G8B8A8 \_ Синт
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>\_Формат DXGI \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>\_Формат DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> \_Функция неточного типа использует инструкции шейдера, которые не имеют достаточно большой точности для получения точного ответа. Альтернативная функция использует таблицу подстановки, хранящуюся в шейдере, чтобы обеспечить точное преобразование с плавающей запятой SRGB->.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>\_Формат DXGI \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>\_Формат DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> \_Функция неточного типа использует инструкции шейдера, которые не имеют достаточно большой точности для получения точного ответа. Альтернативная функция использует таблицу подстановки, хранящуюся в шейдере, чтобы обеспечить точное преобразование с плавающей запятой SRGB->.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>\_Формат DXGI \_ R16G16 \_ float
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>\_Формат DXGI \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>\_Формат DXGI \_ R16G16 \_ uint
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>\_Формат DXGI \_ R16G16 \_ снорм
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Формат DXGI \_ R16G16 \_ Синт
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a>См. также

[Руководство по программированию для HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>См. также

<dl> <dt>

[Руководство по программированию для HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




