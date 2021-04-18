---
title: Структура CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры байт-кода шейдера D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Структура CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713503"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>\_ \_ Структура байта ШЕЙДЕРа CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ байт- \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Байт-код шейдера CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ байт-кода шейдера CD3DX12 \_ .

</dd> <dt>

**явный \_ байт-код шейдера CD3DX12 \_ (const D3D12, \_ байтовый код шейдера \_ &o)**
</dt> <dd>

Создает новый экземпляр \_ байт-кода шейдера CD3DX12 \_ , инициализированного с содержимым другой структуры [**байт- \_ \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**\_Байт-код шейдера CD3DX12 \_ (ID3DBlob \* пшадерблоб)**
</dt> <dd>

Создает новый экземпляр \_ байт-кода шейдера CD3DX12 \_ , инициализируя следующие параметры:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* пшадерблоб

</dd> <dt>

**\_Байт-код шейдера CD3DX12 \_ (const void \* \_ Пшадербитекоде, Size \_ T битекоделенгс)**
</dt> <dd>

Создает новый экземпляр \_ байт-кода шейдера CD3DX12 \_ , инициализируя следующие параметры:

void \* \_ пшадербитекоде

РАЗМЕР \_ T битекоделенгс

</dd> <dt>

**D3D12-байта оператора const константы \_ шейдера \_& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Байтовый код шейдера D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

