---
title: Структура D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Указывает состояние устройства.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8087f45ad94fe3e45f78a1be9d86b30f6f7e3f2c9161b9c4498865b12582436e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124939"
---
# <a name="d3dx11_state_block_mask-structure"></a>\_ \_ Структура маски блока D3DX11 State \_

Указывает состояние устройства.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a>Члены

<dl> <dt>

**ЛИНЕЙЧАТ**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние шейдера вершин.

</dd> <dt>

**вссамплерс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив образцов шейдера вершин. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.

</dd> <dt>

**всшадерресаурцес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив ресурсов шейдера вершин. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.

</dd> <dt>

**всконстантбуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив константных буферов вершинного шейдера. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.

</dd> <dt>

**всинтерфацес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив интерфейсов вершинного шейдера. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.

</dd> <dt>

**HS**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние шейдера поверхности.

</dd> <dt>

**хссамплерс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив образцов поверхности-шейдеров. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.

</dd> <dt>

**хсшадерресаурцес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив ресурсов поверхности-шейдеров. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.

</dd> <dt>

**хсконстантбуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив константных буферов поверхности-шейдеров. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.

</dd> <dt>

**хсинтерфацес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив интерфейсов поверхности-шейдеров. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.

</dd> <dt>

**DS**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние шейдера домена.

</dd> <dt>

**дссамплерс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив образцов шейдера домена. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.

</dd> <dt>

**дсшадерресаурцес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив ресурсов шейдера домена. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.

</dd> <dt>

**дсконстантбуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив константных буферов шейдера домена. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один буферный слот.

</dd> <dt>

**дсинтерфацес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив интерфейсов шейдера домена. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.

</dd> <dt>

**GS**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние шейдера Geometry.

</dd> <dt>

**гссамплерс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив образцов шейдеров Geometry. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.

</dd> <dt>

**гсшадерресаурцес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив ресурсов с геометрическим шейдером. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.

</dd> <dt>

**гсконстантбуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив константных буферов с геометрическим шейдером. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один буферный слот.

</dd> <dt>

**гсинтерфацес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив интерфейсов Geometry-Shader. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.

</dd> <dt>

**PS**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние шейдера пикселей.

</dd> <dt>

**пссамплерс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив образцов построителя текстуры. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.

</dd> <dt>

**псшадерресаурцес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив ресурсов растрового шейдера. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.

</dd> <dt>

**псконстантбуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив константных буферов построителя текстуры. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.

</dd> <dt>

**псинтерфацес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив интерфейсов построителя текстуры. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.

</dd> <dt>

**псунордередакцессвиевс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять неупорядоченные представления доступа шейдера пикселей.

</dd> <dt>

**CS**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние шейдера вычислений.

</dd> <dt>

**кссамплерс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив пробных шейдеров COMPUTE. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.

</dd> <dt>

**ксшадерресаурцес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив ресурсов COMPUTE-Shader. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.

</dd> <dt>

**ксконстантбуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив константных буферов COMPUTE-Shader. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.

</dd> <dt>

**ксинтерфацес**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив интерфейсов COMPUTE-Shader. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.

</dd> <dt>

**ксунордередакцессвиевс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять неупорядоченные представления доступа "вычисление шейдеров".

</dd> <dt>

**иавертексбуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Массив буферов вершин. Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.

</dd> <dt>

**иаиндексбуффер**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние буфера индекса.

</dd> <dt>

**иаинпутлайаут**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние макета входных данных.

</dd> <dt>

**иапримитиветопологи**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние простой топологии.

</dd> <dt>

**омрендертаржетс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояния целевых объектов рендеринга.

</dd> <dt>

**омдепсстенЦилстате**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние шаблона глубины.

</dd> <dt>

**омблендстате**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние смешения.

</dd> <dt>

**рсвиевпортс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояния окна просмотра.

</dd> <dt>

**рссЦиссорректс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояния прямоугольных прямоугольников.

</dd> <dt>

**рсрастеризерстате**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние средства программной прорисовки.

</dd> <dt>

**собуфферс**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояния буферов потоковой передачи.

</dd> <dt>

**Предикация**
</dt> <dd>

Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Логическое значение, указывающее, следует ли сохранять состояние затенения.

</dd> </dl>

## <a name="remarks"></a>Remarks

Маска блока состояния указывает на то, что устройство изменило метод передачи или приема.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

