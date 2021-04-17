---
title: Структура CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры корневого \_ параметра D3D12.
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Структура CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713504"
---
# <a name="cd3dx12_root_parameter-structure"></a>\_Структура корневого \_ параметра CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ корневого \_ параметра D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Параметр CD3DX12 root \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ параметра CD3DX12 root \_ .

</dd> <dt>

**явный \_ параметр CD3DX12 root \_ (const D3D12 \_ корневой \_ параметр &o)**
</dt> <dd>

Создает новый экземпляр \_ корневого \_ параметра CD3DX12, инициализируемый с помощью содержимого другой структуры [**\_ корневого \_ параметра D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

</dd> <dt>

**static Inline Инитасдескриптортабле (D3D12 \_ root \_ Parameter &РУТПАРАМ, uint нумдескрипторранжес, const D3D12 \_ , диапазон дескрипторов \_ \* пдескрипторранжес, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам

UINT Нумдескрипторранжес

[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \*

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасконстантс (D3D12 \_ root \_ Parameter &РУТПАРАМ, uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, видимость D3D12 \_ шейдера видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам

UINT num32BitValues

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасконстантбуффервиев (D3D12 \_ root, \_ параметр &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимость \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасшадерресаурцевиев (D3D12 \_ root, \_ параметр &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимость \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасунордередакцессвиев (D3D12 \_ root, \_ параметр &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимость \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасдескриптортабле (UINT Нумдескрипторранжес, const D3D12 \_ \_ диапазон дескрипторов \* ПДЕСКРИПТОРРАНЖЕС, \_ видимость D3D12 шейдера видимости \_ = D3D12 \_ \_ видимость шейдера \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Нумдескрипторранжес

[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \*

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасконстантс (UINT num32BitValues, UINT Шадеррегистер, UINT Регистерспаце = 0, видимость D3D12 \_ шейдер видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT num32BitValues

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасконстантбуффервиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасшадерресаурцевиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасунордередакцессвиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

участие UINT Регистерспаце = 0

участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Корневой \_ параметр D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





